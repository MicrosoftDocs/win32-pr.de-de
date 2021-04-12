---
title: IMsRdpDeviceCollection2 redirectnow-Methode
description: Erzwingt das umgeleitet oder Entfernen von Geräten, die in der Sammlung ausgewählt oder nicht ausgewählt wurden.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Redirectnow-Methode Remotedesktopdienste
- Redirectnow-Methode Remotedesktopdienste, IMsRdpDeviceCollection2-Schnittstelle
- IMsRdpDeviceCollection2-Schnittstelle Remotedesktopdienste, redirectnow-Methode
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949431"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a>IMsRdpDeviceCollection2:: redirectnow-Methode

Erzwingt das umgeleitet oder Entfernen von Geräten, die in der Sammlung ausgewählt oder nicht ausgewählt wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ in\]
</dt> <dd>

Type: **[ **redirectdevicetype**](redirectdevicetype.md)**

Ein Wert der [**redirectdevicetype**](redirectdevicetype.md) -Enumeration, der den Gerätetyp angibt, der umgeleitet werden soll.

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

 

 





