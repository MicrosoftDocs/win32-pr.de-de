---
description: Ruft alle einem Gerät zugeordneten Scanprofile ab.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: IScanProfileMgr::GetProfilesforDeviceID-Methode (Scanprofilemgr.h)
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
ms.openlocfilehash: 8ca150d02aff2f84becf8b36aca87e2da24b2b83c9ccd85c0cf5a1c5ced0d664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209056"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a>IScanProfileMgr::GetProfilesforDeviceID-Methode

Ruft alle einem Gerät zugeordneten Scanprofile ab.

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

*bstrDeviceID* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die ID des Geräts.

</dd> <dt>

*pulNumProfiles* \[ in, out\]
</dt> <dd>

Typ: **ULONG \***

Wenn sie übergeben wird, ein Zeiger auf die maximale Anzahl von Profilen, die zurückgegeben werden sollen. Wenn zurückgegeben, der ein Zeiger auf die Anzahl der zurückgegebenen Profile ist.

</dd> <dt>

*ppScanProfile* \[ out\]
</dt> <dd>

Typ: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Die Adresse eines Zeigers auf ein Array von Profilen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn die Gesamtzahl der profile, die dem Gerät zugeordnet sind, kleiner als der An *pulNumProfiles* übergebene Wert ist, gibt *pulNumProfiles* diese Summe zurück. Andernfalls wird der gleiche Wert zurückgegeben, der an ihn übergeben wurde.

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

 

 




