---
title: IMsRdpDeviceCollection2 RedirectNow-Methode
description: Erzwingt, dass Geräte, die in der Sammlung ausgewählt oder deaktiviert wurden, umgeleitet oder entfernt werden.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- RedirectNow-Remotedesktopdienste
- RedirectNow-Remotedesktopdienste , IMsRdpDeviceCollection2-Schnittstelle
- IMsRdpDeviceCollection2-Schnittstelle Remotedesktopdienste , RedirectNow-Methode
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
ms.openlocfilehash: 60c92eff142305e95a71c69cdce9789b0d2316e3d5e60b703a7c1aa8e835688f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058918"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a>IMsRdpDeviceCollection2::RedirectNow-Methode

Erzwingt, dass Geräte, die in der Sammlung ausgewählt oder deaktiviert wurden, umgeleitet oder entfernt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ In\]
</dt> <dd>

Typ: **[ **RedirectDeviceType**](redirectdevicetype.md)**

Ein Wert der [**RedirectDeviceType-Enumeration,**](redirectdevicetype.md) der den Typ des geräts angibt, das umgeleitet werden soll.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





