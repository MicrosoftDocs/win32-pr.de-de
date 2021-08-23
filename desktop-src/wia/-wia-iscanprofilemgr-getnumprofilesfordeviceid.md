---
description: Ruft die Anzahl der Scanprofile für das Gerät ab.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: IScanProfileMgr::GetNumProfilesforDeviceID-Methode (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c2af1e4bc73afee090d947e6bcca0060521cb15cf2faff06be8c9a893534ea4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264390"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a>IScanProfileMgr::GetNumProfilesforDeviceID-Methode

Ruft die Anzahl der Scanprofile für das Gerät ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrDeviceID* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die ID des Geräts.

</dd> <dt>

*pulNumProfiles* \[ out\]
</dt> <dd>

Typ: **ULONG \***

Ein Zeiger auf die Anzahl der für das Gerät verfügbaren Profile.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Scan Profile Schema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




