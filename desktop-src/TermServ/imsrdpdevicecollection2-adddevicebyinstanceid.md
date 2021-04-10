---
title: IMsRdpDeviceCollection2 adddevicebyinstanceid-Methode
description: Fügt der Geräte Sammlung ein nicht aufgeführtes Gerät hinzu.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Adddevicebyinstanceid-Methode Remotedesktopdienste
- Adddevicebyinstanceid-Methode Remotedesktopdienste, IMsRdpDeviceCollection2-Schnittstelle
- IMsRdpDeviceCollection2 Interface Remotedesktopdienste, adddevicebyinstanceid-Methode
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
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040124"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a>IMsRdpDeviceCollection2:: adddevicebyinstanceid-Methode

Fügt der Geräte Sammlung ein nicht aufgeführtes Gerät hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ in\]
</dt> <dd>

Type: **[ **redirectdevicetype**](redirectdevicetype.md)**

Ein Wert der [**redirectdevicetype**](redirectdevicetype.md) -Enumeration, der den Typ des hinzugefügten Geräts angibt.

</dd> <dt>

*InstanceId* \[ in\]
</dt> <dd>

Typ: **BSTR**

Der Instanzbezeichner des hinzu zufügenden Geräts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Redirectde vicetype**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





