---
description: Ruft alle einem Gerät zugeordneten Scan Profile ab.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'Iscanprofilemgr:: getprofilesfordeviceid-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349051"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a>Iscanprofilemgr:: getprofilesfordeviceid-Methode

Ruft alle einem Gerät zugeordneten Scan Profile ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die ID des Geräts.

</dd> <dt>

*pulnumprofiles* \[ in, out\]
</dt> <dd>

Typ: **ulong \** _

Bei Übergabe ein Zeiger auf die maximale Anzahl von Profilen, die zurückgegeben werden sollen. Wenn die Rückgabe zurückgegeben wird, ist dies ein Zeiger auf die Anzahl der zurückgegebenen Profile.

</dd> <dt>

_ppScanProfile * \[ out\]
</dt> <dd>

Typ: **[ **iscanprofile**](-wia-iscanprofile.md)\*\***

Die Adresse eines Zeigers auf ein Array von Profilen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die Gesamtanzahl der Profile, die dem Gerät zugeordnet sind, kleiner ist als der an *pulnumprofiles* weiter gegebene Wert, gibt *pulnumprofiles* diese Summe zurück. Andernfalls wird derselbe Wert zurückgegeben, der an ihn übermittelt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscanprofilemgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




