---
description: Gibt die ID des Geräts zurück.
ms.assetid: 72a0843d-36f2-463f-8269-0e91233f1931
title: 'Iscanprofile:: getdeviceid-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetDeviceID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fb0e2597164cb0a82c15cecf394ce7a9e0bec16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344018"
---
# <a name="iscanprofilegetdeviceid-method"></a>Iscanprofile:: getdeviceid-Methode

Gibt die ID des Geräts zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceID(
  [out] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstraude viceid* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **BSTR \** _

Ein Zeiger auf die Geräte-ID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscanprofile**](-wia-iscanprofile.md)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




